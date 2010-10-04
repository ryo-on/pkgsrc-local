# $NetBSD$
#

DISTNAME=	miama
PKGNAME=	${DISTNAME}-1
CATEGORIES=	fonts
MASTER_SITES=	http://github.com/downloads/ryo-on/pkgsrc-local/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://www.dafont.com/miama.font
COMMENT=	cursive font
LICENSE=	open-font-license

PKG_DESTDIR_SUPPORT=	user-destdir

USE_X11BASE=	yes
NO_CONFIGURE=	yes
NO_BUILD=	yes

DOCSDIR=	${PREFIX}/share/doc/${PKGBASE}

INSTALLATION_DIRS=	lib/X11/fonts/TTF \
			${DOCSDIR}

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALL_FONTS=	Miama.ttf

USE_LANGUAGES=	# none

WRKSRC=	${WRKDIR}

do-install:
.for fontfile in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${fontfile} ${DESTDIR}${FONTDIR}
.endfor

.include "../../mk/bsd.pkg.mk"
