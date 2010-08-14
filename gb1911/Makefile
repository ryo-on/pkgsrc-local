# $NetBSD$
#

DISTNAME=	gb1911-2010.07.03
PKGNAME=	${DISTNAME:S/.//g}
CATEGORIES=	fonts
MASTER_SITES=	http://sortsmill.googlecode.com/files/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://crudfactory.com/cf3/gb1911.xhtml
COMMENT=	Goudy Bookletter 1911 font
LICENSE=	public-domain

PKG_DESTDIR_SUPPORT=	user-destdir

WRKSRC=		${WRKDIR}
USE_LANGUAGES=	# none
USE_X11BASE=	YES
NO_BUILD=	YES

DOCSDIR=	${PREFIX}/share/doc/${PKGBASE}

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALLATION_DIRS=	lib/X11/fonts/TTF \
			${DOCSDIR}

INSTALL_FONTS=	GoudyBookletter1911TT.ttf \
		GoudyBookletter1911.otf
INSTALL_DOCS=	COPYING

do-install:
.for filename in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${filename} ${DESTDIR}${FONTDIR}
.endfor
	${INSTALL_DATA} ${WRKSRC}/${INSTALL_DOCS} ${DESTDIR}${DOCSDIR}

.include "../../mk/bsd.pkg.mk"
