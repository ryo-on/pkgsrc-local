# $NetBSD$
#

DISTNAME=	goudy-3.1
CATEGORIES=	fonts
MASTER_SITES=	http://sortsmill.googlecode.com/files/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://sortsmill.googlecode.com/files/
COMMENT=	Sorts Mill Goudy Oldstyle and Italic fonts
LICENSE=	mit

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

INSTALL_FONTS=	GoudyStM.otf GoudyStMTT.ttf \
		GoudyStM-Italic.otf GoudyStMTT-Italic.ttf
INSTALL_DOCS=	COPYING

do-install:
.for filename in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${filename} ${DESTDIR}${FONTDIR}
.endfor
	${INSTALL_DATA} ${WRKSRC}/${INSTALL_DOCS} ${DESTDIR}${FONTDIR}

.include "../../mk/bsd.pkg.mk"
