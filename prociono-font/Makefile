# $NetBSD$
#

DISTNAME=	prociono-2.3
CATEGORIES=	fonts
MASTER_SITES=	http://sortsmill.googlecode.com/files/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://crudfactory.com/cf3/prociono.xhtml
COMMENT=	Prociono font
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

INSTALL_FONTS=	Prociono.otf \
		ProcionoTT.ttf
INSTALL_DOCS=	COPYING

do-install:
.for filename in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${filename} ${DESTDIR}${FONTDIR}
.endfor
	${INSTALL_DATA} ${WRKSRC}/${INSTALL_DOCS} ${DESTDIR}${DOCSDIR}

.include "../../mk/bsd.pkg.mk"
